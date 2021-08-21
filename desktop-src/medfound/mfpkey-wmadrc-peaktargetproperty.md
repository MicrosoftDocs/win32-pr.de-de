---
description: Gibt die gewünschte maximale Lautstärke des Ausgabeaudioinhalts an.
ms.assetid: 231b7296-ca80-4918-bae6-674b976db24c
title: MFPKEY_WMADRC_PEAKTARGET-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79f54d15978bb3f6a34c015886d2aeb2a8ec48a0069669e81ea40bbd79353902
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973229"
---
# <a name="mfpkey_wmadrc_peaktarget-property"></a>MFPKEY \_ WMADRC \_ PEAKTARGET-Eigenschaft

Gibt die gewünschte maximale Lautstärke des Ausgabeaudioinhalts an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszWMADRCPeakTarget

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

Siehe Hinweise.

## <a name="remarks"></a>Hinweise

Sie können diesen Wert für den Decoder zum Zweck der dynamischen Bereichssteuerung festlegen. Er hat jedoch nur dann Auswirkungen, wenn die [ \_ MFPKEY WFPC \_ DRCMODE-Eigenschaft](mfpkey-wmadec-drcmodeproperty.md) festgelegt ist.

Wenn Sie eine dynamische Bereichssteuerung vom Decoder anfordern, wenn diese Eigenschaft nicht festgelegt ist, berechnet der Codec einen Standardwert.

Verwenden Sie [die Eigenschaften MFPKEY \_ WMADRC \_ AVGREF](mfpkey-wmadrc-avgrefproperty.md) und [MFPKEY \_ WMADRC \_ PEAKREF,](mfpkey-wmadrc-peakrefproperty.md) um die entsprechenden Werte für diese Eigenschaft zu berechnen.

Weitere Informationen zur Dynamischen Bereichssteuerung finden Sie im Webartikel [Windows Media Audio Professional Codec Features](/previous-versions/ms867218(v=msdn.10)).

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

 

 
