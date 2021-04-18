---
description: Gibt Informationen zum Long-Term Reference (LTR)-Frame an und wird im Ausgabe Beispiel zurückgegeben.
ms.assetid: 0632D780-C56B-4FDB-8A76-B7A7DE414242
title: MFSampleExtension_LongTermReferenceFrameInfo-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3af85ffa5876cdf58a21a6933c46f460c23e7456
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106354281"
---
# <a name="mfsampleextension_longtermreferenceframeinfo-attribute"></a>Mfsampleextension \_ longtermreferenceframeinfo-Attribut

Gibt Informationen zum Long-Term Reference (LTR)-Frame an und wird im Ausgabe Beispiel zurückgegeben.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

**H. 264/AVC-Encoder:**

Encoder müssen dieses Attribut für das Ausgabe Beispiel zurückgeben, wenn die Anwendung die Ltr-Frames steuert, die von [codecapi \_ avencvideoltrbuffercontrol](codecapi-avencvideoltrbuffercontrol.md)angegeben werden.

Mfsampleextension \_ longtermreferenceframeinfo gibt bis zu zwei Felder zurück.

Das erste Feld (Bits \[ 0.. 15) \] ist *longtermframeidx* , das dem Ausgabe Frame zugeordnet ist, wenn er als Ltr-Frame markiert ist. Der erste Wert ist 0xFFFF, wenn dieser Ausgabe Rahmen ein kurzfristiger Verweis Rahmen oder ein nicht Verweis Rahmen ist.

Das zweite Feld, Bits \[ 16.. 31 \] , ist eine Bitmap, die aus " *maxnumltrframes* " zahlreiche Bits besteht, die angeben, welche Ltr-Frames zum Codieren dieses Ausgabe Frames verwendet wurden, beginnend bei Bit 16. Der Rest der Bits muss auf 0 festgelegt werden. Der zweite Wert ist 0, wenn dieser Ausgabe Rahmen nicht mithilfe von Ltr-Frames codiert wird. *Maxnumltrframes* ist die maximale Anzahl von Ltr-Frames, die über [codecapi \_ avencvideoltrbuffercontrol](codecapi-avencvideoltrbuffercontrol.md)festgelegt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1 \[ Desktop-Apps \| UWP-apps\]<br/>                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




