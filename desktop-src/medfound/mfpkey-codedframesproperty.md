---
description: Gibt die Anzahl von Videoframes an, die vom Codec codiert werden.
ms.assetid: 4a812609-137f-4f7f-aa55-89e26d7f1972
title: MFPKEY_CODEDFRAMES-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e836f2177311a2ffc13065187a1affce93c6dbe74ff9ff4c99ef78a6f492b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954730"
---
# <a name="mfpkey_codedframes-property"></a>MFPKEY \_ CODEDFRAMES-Eigenschaft

Gibt die Anzahl von Videoframes an, die vom Codec codiert werden.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszWMVCCodedFrames

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="remarks"></a>Hinweise

Dieser Wert entspricht [MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md) abzüglich der Frames, die aufgrund von Einschränkungen der Bitrate gelöscht wurden. Sie können diesen Wert erhalten, nachdem Sie die Beispiele übergeben haben.

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

 

 




