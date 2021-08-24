---
description: Gibt die Spitzenbitrate in Bits pro Sekunde an, die für die eingeschränkte VBR-Wiedergabe (Variable-Bit-Rate) mit 2 Durchgang verwendet wird.
ms.assetid: 51f161d2-f832-48d5-8f16-861e2a98a7f7
title: MFPKEY_RMAX-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e80f679d0ed1213a54a4f22bc5d8bfc79f41b93fa05c446c8b6ed0f589183b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119398400"
---
# <a name="mfpkey_rmax-property"></a>MFPKEY \_ RMAX-Eigenschaft

Gibt die Spitzenbitrate in Bits pro Sekunde an, die für die eingeschränkte VBR-Wiedergabe (Variable-Bit-Rate) mit 2 Durchgang verwendet wird.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszWMVCMaxBitrate

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

Keine Standardeinstellung.

## <a name="remarks"></a>Hinweise

Dieser Wert stellt die Spitzenbitrate für die Wiedergabe dar. Der Wert [von MFPKEY \_ BMAX](mfpkey-bmaxproperty.md) wird verwendet, um den Puffer in Bezug auf diese Bitrate zu beschreiben. Tatsächlich ähnelt die eingeschränkte VBR der konstanten Bitrate (CBR), die diesen Wert als Bitrate verwendet. Ein eingeschränkter VBR-Stream kann jedoch mit einer niedrigeren Bitrate abgespielt werden, solange der Puffer erhöht wird.

Sie müssen diesen Wert für die VBR-Codierung mit zwei Durchgangsspitzen festlegen. Nachdem Sie mit der Verarbeitung von Beispielen begonnen haben, dürfen Sie diesen Wert erst abfragen, wenn Sie die Codierung des Streams abgeschlossen haben. Der Encoder interpretiert eine Anforderung für diesen Wert als Signal, dass die Codierungssitzung beendet ist. Das nächste Beispiel, das Sie verarbeiten, wird als Anfang einer neuen Sitzung behandelt.

In der Regel ist dieser Wert zwei- bis dreimal größer als der Wert von [MFPKEY \_ RAVG](mfpkey-ravgproperty.md).

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

 

 




