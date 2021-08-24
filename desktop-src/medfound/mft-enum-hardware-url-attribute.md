---
description: Enthält die symbolische Verknüpfung für eine hardwarebasierte Media Foundation Transform (MFT).
ms.assetid: 7e153051-a167-4ff7-8178-b290d8a1345e
title: MFT_ENUM_HARDWARE_URL_Attribute -Attribut (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7119ea4bde7900087f706cb6fbc77c845721debab54dfa05b48f5c0094b1e29e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722585"
---
# <a name="mft_enum_hardware_url_attribute-attribute"></a>Attribut des \_ MFT-ENUM-HARDWARE-URL-Attributs \_ \_ \_

Enthält die symbolische Verknüpfung für eine hardwarebasierte Media Foundation Transform (MFT).

## <a name="data-type"></a>Datentyp

**Wchar\***

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DEN ATTRIBUTEAttributes::GetString auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)

Rufen Sie ZUM Festlegen dieses [**Attributs DEN WERTATTRIBUTEs::SetString auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)

## <a name="remarks"></a>Hinweise

Dieses Attribut wird von hardwarebasierten MFTs unterstützt. Der Wert des Attributs ist die symbolische Verknüpfung für den Gerätetreiber. Dieses Attribut wird auch für die VON der [**MFTEnumEx-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) zugeordneten [**ATTRIBUTActivate-Zeiger**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) festgelegt, wenn diese Zeiger hardwarebasierte MFTs darstellen.

Die symbolische Verknüpfung sollte als nicht transparente Zeichenfolge betrachtet werden. Fragen Sie das [MFT \_ FRIENDLY \_ NAME-Attribut](mft-friendly-name-attribute.md) ab, um den Anzeigenamen für ein Gerät zu erhalten.

Für Software-MFTs sollte dieses Attribut nicht festgelegt sein.

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

[Hardware-MFTs](hardware-mfts.md)
</dt> <dt>

[Transformieren von Attributen](transform-attributes.md)
</dt> </dl>

 

 




