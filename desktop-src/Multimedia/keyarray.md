---
title: Keyarray (MMSYSTEM. h)
description: Keyarray gibt einen Typ an, der verwendet wird, um ein Array von Schlüsseln zu definieren.
ms.assetid: af1a1d2f-4558-4374-93ab-5a705fc879ca
keywords:
- keyarray midipatchsize
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6e45e46417fb3b6653ecae605aa60f775c1d654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346716"
---
# <a name="keyarray"></a>Keyarray

Keyarray gibt einen Typ an, der verwendet wird, um ein Array von Schlüsseln zu definieren.


```C++
typedef WORD KEYARRAY[MIDIPATCHSIZE];
```



<dl> <dt>

**keyarray \[ midipatchsize\]**
</dt> <dd>

Jedes Element im Array entspricht einem Key-basierten Percussion-Patch, wobei jede der 16 Bits einen der 16 MIDI-Kanäle darstellt. Bits werden für jeden der Kanäle festgelegt, die diesen bestimmten Patch verwenden. Wenn beispielsweise der Percussion-Patch für die Schlüsselnummer 60 von den physischen MIDI-Kanälen 9 und 15 verwendet wird, sollte das Element 60 des Arrays auf 0x8200 festgelegt werden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Version<br/>                  | Digital Instrumentation Digital Interface (MIDI), MIDI-Typen<br/>                                        |
| Header<br/>                   | <dl> <dt>MMSYSTEM. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MIDI-Typen](midi-event-types.md)
</dt> </dl>

 

 





