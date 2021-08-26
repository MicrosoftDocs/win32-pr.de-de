---
description: Gibt die Anzahl der Threads an, die vom Encoder verwendet werden.
ms.assetid: 2f463cba-2512-455d-9ce1-8797682d4d67
title: MFPKEY_NUMTHREADS-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ac8b6ec040ba07a2e38b1e9d8e2df6cf0fcbfcdbba14481e9b50379ecc10df5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953910"
---
# <a name="mfpkey_numthreads-property"></a>MFPKEY \_ NUMTHREADS-Eigenschaft

Gibt die Anzahl der Threads an, die vom Encoder verwendet werden.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszWMVCNumThreads

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

1

## <a name="remarks"></a>Hinweise

Dieser Wert soll die Codierung in mehrere Threads unterteilen, um Computer mit mehreren Prozessoren zu nutzen. Das Aufteilen von Codierungsaufgaben in mehrere Threads kann im Vergleich zu einem einzelnen Thread zu einem geringfügigen Qualitätsverlust führen.

Für den Videoencoder (wmvencod.dll), der mit Windows XP und Windows Vista veröffentlicht wurde, sollte diese Eigenschaft auf 1, 2 oder 4 festgelegt werden. Andere Werte werden abgerundet.

Für den Videoencoder (wmvencod.dll), der mit Windows 7 veröffentlicht wurde, sollte diese Eigenschaft auf 1, 2, 4 oder 8 festgelegt werden. Andere Werte werden abgerundet.

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

 

 




