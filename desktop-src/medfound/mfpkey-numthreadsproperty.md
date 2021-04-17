---
description: Gibt die Anzahl der Threads an, die vom Encoder verwendet werden.
ms.assetid: 2f463cba-2512-455d-9ce1-8797682d4d67
title: MFPKEY_NUMTHREADS-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c93f6d38e3bb79bbb692f9bec1b1dc0edb232d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528664"
---
# <a name="mfpkey_numthreads-property"></a>Mfpkey- \_ numThreads (Eigenschaft)

Gibt die Anzahl der Threads an, die vom Encoder verwendet werden.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmvcnumthreads

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

1

## <a name="remarks"></a>Bemerkungen

Dieser Wert soll die Codierung in mehrere Threads aufteilen, um die Vorteile von Computern mit mehreren Prozessoren zu nutzen. Wenn Codierungs Aufgaben in mehrere Threads aufgeteilt werden, kann dies zu einer geringfügigen Abnahme der Qualität im Vergleich zu einem einzelnen Thread führen.

Für den Video Encoder (wmvencod.dll), der mit Windows XP und Windows Vista veröffentlicht wurde, sollte diese Eigenschaft auf 1, 2 oder 4 festgelegt werden. Andere Werte werden abgerundet.

Für den Video Encoder (wmvencod.dll), der mit Windows 7 veröffentlicht wurde, sollte diese Eigenschaft auf 1, 2, 4 oder 8 festgelegt werden. Andere Werte werden abgerundet.

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

 

 




