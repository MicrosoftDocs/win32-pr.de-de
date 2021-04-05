---
description: Gibt die Inhalts Teile an, die vom Voice-Codec als Musik codiert werden sollen.
ms.assetid: c63034ce-33d7-4f2f-9498-fc16e25b6d4d
title: MFPKEY_WMAVOICE_ENC_EDL-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f3ac85ebd3a0542fbcf6554205d0b2f2623957c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755305"
---
# <a name="mfpkey_wmavoice_enc_edl-property"></a>Mfpkey \_ wmavoice \_ ENC \_ EDL (Eigenschaft)

Gibt die Inhalts Teile an, die vom Voice-Codec als Musik codiert werden sollen.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmacvoicebuffer

## <a name="data-type"></a>Datentyp

VT \_ BSTR

## <a name="default-value"></a>Standardwert

Für dieses Feld gibt es keinen Standardwert. Wenn diese Eigenschaft nicht festgelegt ist, verwendet der Codec den Wert der Eigenschaft [mfpkey \_ wmavoice \_ ENC \_ musicvoiceclassmode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) , um zu bestimmen, wie der Inhalt codiert werden soll.

## <a name="remarks"></a>Bemerkungen

Sie können diese Eigenschaft verwenden, wenn der automatische Modus des Codecs keine zufriedenstellenden Ergebnisse liefert.

Dieser Wert ist eine durch Trennzeichen getrennte Zeichenfolge, die mindestens vier ganze Zahlen enthält. Die erste ganze Zahl ist die Versionsnummer. Verwenden Sie für diesen Wert immer 1. Die zweite Ganzzahl ist die Anzahl der Abschnitte, die als Musik codiert werden müssen. Die zweite Ganzzahl ist eine Reihe von Werten, die Bereiche in Millisekunden darstellen, ein paar für jeden Inhalts Abschnitt, der als Musik codiert werden muss.

"1, 2100200500600" informiert den Encoder beispielsweise über die Verwendung von Version 1 mit 2 Teilen der Musik. Der erste Musik Abschnitt beginnt bei 100 MS und endet um 200 ms. Der zweite Musik Abschnitt beginnt bei 500 ms und endet um 600 ms.

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

 

 




