---
description: Gibt den Modus des voicecodec an.
ms.assetid: 8425cdab-e43c-41ca-9c20-09ab6a5f06f4
title: MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9776c76f2a8863afe73626f5a2940de2c0ccb7cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345204"
---
# <a name="mfpkey_wmavoice_enc_musicspeechclassmode-property"></a>Mfpkey \_ wmavoice \_ ENC \_ musicvoiceclassmode (Eigenschaft)

Gibt den Modus des voicecodec an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmacmusicredner classmode

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

1

## <a name="remarks"></a>Bemerkungen

Mit dem Wert 1 wird dem Codec mitgeteilt, dass der Inhalt sprach geschützt ist, bei einem Wert von 2 der Codec den Modus automatisch bestimmt, und jeder andere Wert informiert den Codec über die Verwendung des Musik Modus.

Wenn der automatische Modus gemischte Sprache und Musik nicht ordnungsgemäß codiert, können Sie mithilfe der Eigenschaft [mfpkey \_ wmavoice \_ ENC \_ EDL](mfpkey-wmavoice-enc-edlproperty.md) die Codierung für einzelne Abschnitte der Datei angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




