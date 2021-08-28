---
description: Gibt den Modus des Sprachcodecs an.
ms.assetid: 8425cdab-e43c-41ca-9c20-09ab6a5f06f4
title: MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303a86adbf9c443149ff78a47d19922284e38d2c0aeb56dcc13a74ca20cd54a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113120"
---
# <a name="mfpkey_wmavoice_enc_musicspeechclassmode-property"></a>MFPKEY \_ WMAVOICE \_ ENC \_ MusicSpeechClassMode-Eigenschaft

Gibt den Modus des Sprachcodecs an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszWMACModeSpeechClassMode

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

1

## <a name="remarks"></a>Hinweise

Der Wert 1 informiert den Codec darüber, dass der Inhalt sprachgeeigent ist. Bei einem Wert von 2 wird der Modus automatisch vom Codec bestimmt, und jeder andere Wert informiert den Codec über die Verwendung des Musikmodus.

Wenn der automatische Modus Mixed Voice und Musik nicht ordnungsgemäß codiert, können Sie die Codierung für einzelne Abschnitte der Datei mithilfe der [MFPKEY \_ WMAVOICE \_ ENC \_ EDL-Eigenschaft](mfpkey-wmavoice-enc-edlproperty.md) angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 




