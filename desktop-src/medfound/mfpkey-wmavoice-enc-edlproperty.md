---
description: Gibt die Teile des Inhalts an, die vom Sprachcodec als Musik codiert werden sollen.
ms.assetid: c63034ce-33d7-4f2f-9498-fc16e25b6d4d
title: MFPKEY_WMAVOICE_ENC_EDL-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ffc9f68c7122897c9f5032e9ac0e4fc93c596b5ce65f18d44fb6af6dff2dd2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713720"
---
# <a name="mfpkey_wmavoice_enc_edl-property"></a>MFPKEY \_ WMAVOICE \_ ENC \_ EDL-Eigenschaft

Gibt die Teile des Inhalts an, die vom Sprachcodec als Musik codiert werden sollen.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszWMACVoiceBuffer

## <a name="data-type"></a>Datentyp

VT \_ BSTR

## <a name="default-value"></a>Standardwert

Für dieses Feld gibt es keinen Standardwert. Wenn diese Eigenschaft nicht festgelegt ist, verwendet der Codec den Wert der [MFPKEY \_ WMAVOICE \_ ENC \_ MusicSpeechClassMode-Eigenschaft,](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) um zu bestimmen, wie der Inhalt codiert werden soll.

## <a name="remarks"></a>Hinweise

Sie können diese Eigenschaft verwenden, wenn der automatische Modus des Codecs keine zufriedenstellenden Ergebnisse liefert.

Dieser Wert ist eine durch Trennzeichen getrennte Zeichenfolge, die mindestens vier ganze Zahlen enthält. Die erste ganze Zahl ist die Versionsnummer. Verwenden Sie immer 1 für diesen Wert. Die zweite ganze Zahl ist die Anzahl der Abschnitte, die als Musik codiert werden müssen. Nach der zweiten ganzen Zahl folgen mehrere Wertepaare, die Bereiche in Millisekunden darstellen, ein Paar für jeden Abschnitt des Inhalts, der als Musik codiert werden muss.

Beispielsweise informiert "1,2,100,200,500,600" den Encoder, Version 1 mit zwei Musikabschnitten zu verwenden. Der erste Musikabschnitt beginnt bei 100 ms und endet bei 200 ms. Der zweite Musikabschnitt beginnt bei 500 ms und endet bei 600 ms.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 




