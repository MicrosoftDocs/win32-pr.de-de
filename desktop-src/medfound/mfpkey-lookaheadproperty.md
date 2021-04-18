---
description: Gibt die Anzahl der Frames nach dem aktuellen Frame an, den der Codec vor dem Codieren des aktuellen Frames auswerten soll.
ms.assetid: e5cdd066-e25a-4107-9523-5611bd792372
title: MFPKEY_LOOKAHEAD-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1a024c4d0be6ef7ab16c4bf51f290b01de3282b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354638"
---
# <a name="mfpkey_lookahead-property"></a>Mfpkey- \_ Lookahead-Eigenschaft

Gibt die Anzahl der Frames nach dem aktuellen Frame an, den der Codec vor dem Codieren des aktuellen Frames auswerten soll.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmvclookahead

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

0

## <a name="remarks"></a>Bemerkungen

Wenn der Codec Lookahead verwendet, kann er das Video effizienter codieren.

Das Writer-Objekt des Windows Media Format SDK erwartet, dass der Codec die einzelnen Stichproben sofort codiert. Dies hat zur Folge, dass diese Funktion in Software, die das Writer-Objekt verwendet (einschließlich Windows Media Encoder und Windows Media Player), nicht ordnungsgemäß funktioniert. Alle Dateneinheiten Erweiterungen, die Video Frames zugeordnet sind, werden an den falschen Ausgabe Rahmen angefügt. Die Anzahl der Frames, nach denen die Dateneinheiten Erweiterungen falsch platziert werden, entspricht der Anzahl der verwendeten Frames von Lookahead.

Gültige Lookahead-Werte reichen von 0 bis 16 Frames. Der empfohlene Wert ist 16.

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

 

 




