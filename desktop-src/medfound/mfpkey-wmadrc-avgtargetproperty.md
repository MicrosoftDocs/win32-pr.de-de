---
description: Gibt die gewünschte durchschnittliche Lautstärke des Audioausgabeinhalts an.
ms.assetid: 2e59537f-ee14-4186-b312-297225e91120
title: MFPKEY_WMADRC_AVGTARGET-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c1cdd3143d7ca91be3856c9eaf3b7daecbfd80bff53fbd36c20c830dcb64e1d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887610"
---
# <a name="mfpkey_wmadrc_avgtarget-property"></a>MFPKEY \_ WMADRC \_ AVGTARGET-Eigenschaft

Gibt die gewünschte durchschnittliche Lautstärke des Audioausgabeinhalts an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszWMADRCAverageTarget

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

Siehe Hinweise.

## <a name="remarks"></a>Hinweise

Sie können diesen Wert für den Decoder zum Zweck der dynamischen Bereichssteuerung festlegen. Er hat jedoch nur dann Auswirkungen, wenn die [ \_ MFPKEY WFPC \_ DRCMODE-Eigenschaft](mfpkey-wmadec-drcmodeproperty.md) festgelegt ist.

> [!Note]  
> Das Festlegen des durchschnittlichen Zielwerts wird nicht empfohlen. Das Anpassen des Durchschnittswerts wirkt sich nicht auf den Unterschied zwischen lautem und weichem Sound aus. Stattdessen wird das durchschnittliche Gesamtvolumen reduziert oder verstärkt, was zu unerwünschten Verzerrungen während der Wiedergabe führen kann.

 

Wenn Sie eine dynamische Bereichssteuerung vom Decoder anfordern, wenn diese Eigenschaft nicht festgelegt ist, berechnet der Codec einen Standardwert.

Verwenden Sie [die Eigenschaften MFPKEY \_ WMADRC \_ AVGREF](mfpkey-wmadrc-avgrefproperty.md) und [MFPKEY \_ WMADRC \_ PEAKREF,](mfpkey-wmadrc-peakrefproperty.md) um die entsprechenden Werte für diese Eigenschaft zu berechnen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 




