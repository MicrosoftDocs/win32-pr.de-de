---
description: Enthält den Anzeigenamen für eine hardwarebasierte Media Foundation Transformation (MFT).
ms.assetid: 8f2634e8-6bdd-463a-893a-6dc616c8333d
title: MFT_FRIENDLY_NAME_Attribute -Attribut (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b867db021c43679fef026022bf95bda1186a679eb544465393562b0a51d5d7af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554920"
---
# <a name="mft_friendly_name_attribute-attribute"></a>MFT \_ FRIENDLY \_ \_ NAME-Attributattribut

Enthält den Anzeigenamen für eine hardwarebasierte Media Foundation Transformation (MFT).

## <a name="data-type"></a>Datentyp

**Wchar\***

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DEN ATTRIBUTEAttributes::GetString auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)

Rufen Sie ZUM Festlegen dieses [**Attributs DEN WERTATTRIBUTEs::SetString auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)

## <a name="remarks"></a>Hinweise

Dieses Attribut wird von hardwarebasierten MFTs unterstützt. Sie wird auch für die VON der [**MFTEnumEx-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) zugeordneten [**ZEIGER FÜR DIEACTIVate-Funktion**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) festgelegt, wenn diese Zeiger hardwarebasierte MFTs darstellen.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server 2008 \[ \| R2-Desktop-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Transformieren von Attributen](transform-attributes.md)
</dt> </dl>

 

 




