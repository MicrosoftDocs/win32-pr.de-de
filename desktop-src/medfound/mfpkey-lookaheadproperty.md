---
description: Gibt die Anzahl der Frames nach dem aktuellen Frame an, die der Codec vor dem Codieren des aktuellen Frames auswertet.
ms.assetid: e5cdd066-e25a-4107-9523-5611bd792372
title: MFPKEY_LOOKAHEAD-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa5b11abbacc19a4a66dda785d628b1f5d67f636a0f02c7392402ad64a7c3926
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113330"
---
# <a name="mfpkey_lookahead-property"></a>MFPKEY \_ LOOKAHEAD-Eigenschaft

Gibt die Anzahl der Frames nach dem aktuellen Frame an, die der Codec vor dem Codieren des aktuellen Frames auswertet.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszWMVCLookAhead

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

0

## <a name="remarks"></a>Hinweise

Wenn der Codec Lookahead verwendet, kann er das Video effizienter codieren.

Das Writer-Objekt des Windows Media Format SDK erwartet, dass der Codec jedes Beispiel sofort codiert. Daher funktioniert dieses Feature nicht ordnungsgemäß in Software, die das Writer-Objekt verwendet (einschließlich Windows Media Encoder und Windows Media Player). Alle Dateneinheitserweiterungen, die Videoframes zugeordnet sind, werden an den falschen Ausgabeframe angefügt. Die Anzahl der Frames, in denen die Dateneinheitserweiterungen falsch platziert werden, entspricht der Anzahl der verwendeten Lookaheadframes.

Gültige Lookaheadwerte liegen zwischen 0 und 16 Frames. Der empfohlene Wert ist 16.

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

 

 




